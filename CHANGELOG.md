# Next version
- Your contribution!
- Update [README.md](README.md)
- Fix bug when no time entries were to be submitted
- **Breaking change**: Specific days must be configured in the special `specific_days` section in the configuration file
- Specific weeks or months can be defined with `specific_weeks` and `specific_months` configuration
~~~json
assignments:
  default_day:
    - project_id: 1234
      task_id:    100
      hours:      3
    - project_id: 9999
      task_id:    120
      hours:      2
    - project_id: 4321
      task_id:    424
      hours:      2
  specific_days:
    # Quotes around day are mandatory
    # On leave: use an empty array
    '2016-01-17': []
    # Specific day: redefine each tasks
    '2017-12-19':
      - project_id: 1234
        task_id:    456
        hours:      6
      - project_id: 4321
        task_id:    424
        hours:      1
  specific_weeks:
    '2016-52': [] # Christmas week
  specific_months:
    '2016-07': [] # No work on July
~~~

# Version 1.2.0
- Update [README.md](README.md)
- Add `--clear` option to delete time entries
- Fix a typo on Projet URL
- Fix formatting tasks list when mutliple tasks are associated to an assignment

# Version 1.1.0
- Remove `bin/console` from the Gem
- Add a ConfigParser and extract code into models
- Update Gem metadata
- Specify ruby 2.2 as minimum ruby version for the gem
- Add --show option to print TimeEntries registered
- Add --start=2017-01-31 --end=2017-02-10 options for date options. Beware: it includes Saturdays and Sundays

# Version 1.0.0
- Initial release
