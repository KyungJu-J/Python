```python
import logging

logger = logging.getLogger('my_logger')
logger.setLevel(logging.DEBUG)

# 콘솔 출력용 핸들러 추가
ch = logging.StreamHandler()
ch.setLevel(logging.ERROR)
formatter = logging.Formatter("%(asctime)s [%(levelname)s] %(message)s")
ch.setFormatter(formatter)
logger.addHandler(ch)  

# 파일 출력용 핸들러 추가
fh = logging.FileHandler("my_logger.log")
fh.setLevel(logging.DEBUG)
formatter = logging.Formatter("%(asctime)s [%(levelname)s] %(message)s")
fh.setFormatter(formatter)
logger.addHandler(fh)

logger.debug("debug message")
logger.info("info message")
logger.warning("warning message")
logger.error("error message")
logger.critical("critical message")
```
