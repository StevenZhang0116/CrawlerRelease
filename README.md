# crawler_release

An organized and embedded module to scrap information and download pdfs from the ScienceDirect. Supports multithreading works and improves the databases' stability and connectivity (generate unique identifiers to show the state of data). Implements clear and concise APIs and shows understandable outputs. Also, the program is easily extendable to other websites in case of need by modifying the keyword_searcher.py file. Store downloaded PDFs in _cfg.type_blob format

The program's functionalities are listed in the following: 

### help
        show this page.

### show config 
        show config information to run.

### build task <task_id> <keywords_file_path>
        build url list for searching keywords from sciencedirect.com
        params:
                task_id - url list name.
                keywords_file_path - excel file path containing keywords pairs.

### search task <task_id> [max_load_count]
        search sciencedirect.com with urls in task and build 
                info and pdf's address.
        params:
                task_id - url list name.
                max_load_count - optional.max run count,
                        if beyond,stop the process.all tasks by default.

### remove task <task_id>
        remove all task information specified by task_id.
        params:
                task_id - the task id.

### download task <task_id> [max_load_count]
        download pdf file and save into DB.
        params:
                task_id - the task id.
                max_load_count - max run count,all by default.
                        if beyond,the process is stopped.

### sum task
        summary report for tasks.

### sum pdf
        summary report for pdf downloading.

### exp pdf <task=xxx|name=xxx> [...]
        export pdf file from db to hard-drive.you can input some
        conditions such as task,name ext.to search db and export.

