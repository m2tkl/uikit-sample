<template>
  <div>
    <div class="uk-card uk-card-default uk-card-small">
      <div class="uk-card-header">
        <h3 class="uk-card-title">Actions</h3>
      </div>
      <div class="uk-card-body">
        <div class="uk-button-group">
          <div class="uk-flex uk-flex-wrap uk-flex-left">
            <button class="uk-button uk-button-primary uk-button-small">
              <span uk-icon="play"></span>
              Start
            </button>
            <button class="uk-button uk-button-danger uk-button-small">
              <span uk-icon="ban"></span>
              Stop
            </button>
            <button class="uk-button uk-button-danger uk-button-small">
              <span uk-icon="close"></span>
              Kill
            </button>
            <button class="uk-button uk-button-primary uk-button-small">
              <span uk-icon="refresh"></span>
              Restart
            </button>
            <button class="uk-button uk-button-primary uk-button-small">
              <span uk-icon="close"></span>
              Pause
            </button>
            <button class="uk-button uk-button-primary uk-button-small">
              <span uk-icon="play-circle"></span>
              Resume
            </button>
            <button class="uk-button uk-button-primary uk-button-small">
              <span uk-icon="trash"></span>
              Remove
            </button>
          </div>
        </div>
      </div>
    </div>

    <div class="uk-margin">
      <div class="uk-card uk-card-default uk-card-small">
        <div class="uk-card-header">
          <h3 class="uk-card-title">Container status</h3>
        </div>
        <div class="uk-card-body">
          <form class="uk-form-horizontal">
            <div>
              <label class="uk-form-label">ID</label>
              <div class="uk-form-controls">{{ $route.path }}</div>
            </div>
            <hr>
            <div class="uk-margin">
              <label class="uk-form-label">Name</label>
              <div class="uk-form-controls">Hoge</div>
            </div>
            <hr>
            <div class="uk-margin">
              <label class="uk-form-label">Status</label>
              <div class="uk-form-controls">running</div>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>
